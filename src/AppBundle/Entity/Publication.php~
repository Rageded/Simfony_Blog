<?php

namespace AppBundle\Entity;

use Doctrine\ORM\Mapping as ORM;
use Doctrine\Common\Collections\ArrayCollection;

/**
 * Publication
 *
 * @ORM\Table(name="publication")
 * @ORM\Entity(repositoryClass="AppBundle\Repository\PublicationRepository")
 */
class Publication
{


/**
* @var ArrayCollection
*
* @ORM\OneToMany(targetEntity="Issue", mappedBy="publication")
*/

    /**
     * @var int
     *
     * @ORM\Column(name="id", type="integer")
     * @ORM\Id
     * @ORM\GeneratedValue(strategy="AUTO")
     */
    private $id;

    /**
     * @var string
     *
     * @ORM\Column(name="name", type="string", length=255)
     */
    private $name;


    public function __construct(){
        $this->issues = new ArrayCollection();
    }

    /**
     * Get id
     *
     * @return int
     */
    public function getId()
    {
        return $this->id;
    }

    /**
     * Set name
     *
     * @param string $name
     *
     * @return Publication
     */
    public function setName($name)
    {
        $this->name = $name;

        return $this;
    }

    /**
     * Get name
     *
     * @return string
     */
    public function getName()
    {
        return $this->name;
    }

    /**
    * Remove issues
    *
    * @param \AppBundle\Entity\Issue $issue)
    */
    public function removeIssue(\AppBundle\Entity\Issue $issue)
    {
        $this->issue->removeElement($issue);
    }

    /**
    * Get issues
    *
    * @return \Doctrine\Common\Collections\Collection
    */
    public function getIssue()
    {
      return $this->issue;
    }

    /**
    * Render a Publication as a string
    *
    * @return string
    */

    public function __toString(){
      return $this->getName();
    }

}
