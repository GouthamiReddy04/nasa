using System;
using System.Collections.Generic;

class CelestialBody
{
    public string Name { get; }
    public double DistanceFromSun { get; } // Distance in millions of kilometers

    public CelestialBody(string name, double distance)
    {
        Name = name;
        DistanceFromSun = distance;
    }

    public override string ToString()
    {
        return $"{Name} - Distance from Sun: {DistanceFromSun} million km";
    }
}

class Program
{
    static void Main(string[] args)
    {
        // Create celestial bodies
        CelestialBody sun = new CelestialBody("Sun", 0);
        CelestialBody jupiter = new CelestialBody("Jupiter", 778);
        List<CelestialBody> asteroids = new List<CelestialBody>
        {
            new CelestialBody("Asteroid 1", 778.2),
            new CelestialBody("Asteroid 2", 779),
            new CelestialBody("Asteroid 3", 779.5)
        };
        CelestialBody lusiSpacecraft = new CelestialBody("Lusi Spacecraft", 779.8);

        // Display information
        Console.WriteLine("Solar System Simulation");
        Console.WriteLine(sun);
        Console.WriteLine(jupiter);
        foreach (var asteroid in asteroids)
        {
            Console.WriteLine(asteroid);
        }
        Console.WriteLine(lusiSpacecraft);
    }
}
